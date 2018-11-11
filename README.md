### posix-spawn
---
https://github.com/rtomayko/posix-spawn

```
child = POSIX::Spawn::Child.build('git', 'log', :max => 100)
child.exec!
rescue POSIX::Spawn::MaximumOutputExceeded
end
child.out

require 'posix/spawn'
child = POSIX::Spawn::Child.new('it', '--help')

child.out
child.err
child.status

child = POSIX::Spawn::Child.new('bc', :input => '40 + 2')
child.out
```

```ruby
require 'posix/spawn'
pid = POSIX::Spawn::spawn('echo', 'hello world')
stat = Process::waitpid(pid)

require 'posixx/spawn'
class YourGreatClass
  include POSIX::Spawn
  def speak(message)
    pid = spqwn('echo', message)
    Process::waitpid(pid)
  end
  def calculate(expression)
    pid, in, out, err = popen4('bc')
    in.write(expression)
    in.close
    out.read
  ensure
    [in, out, err].each { |io| io.close if !io.closed? }
    Process::waitpid(pid)
  end
end

```

```
```
