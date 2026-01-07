**What is Git?**

- Git is a Version Control System (VCS).
  That means it’s a tool that helps developers track changes in their code, work together, and manage different versions of a project.

**What is GitHub?**

- GitHub is an online platform (a website + service) built on top of Git.
  It’s like a cloud home for your Git repositories.

**Git Command**
<table border="1" cellpadding="10" cellspacing="0" width="100%">
  <thead>
    <tr>
      <th>ক্রমিক</th>
      <th>কমান্ড</th>
      <th>বাংলা ব্যাখ্যা</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td><code>git init</code></td>
      <td>নতুন একটি Git repository তৈরি করে এবং একটি প্রজেক্টকে version control-এর আওতায় আনে।</td>
    </tr>
    <tr>
      <td>2</td>
      <td><code>git status</code></td>
      <td>
        বর্তমান repository-এর ফাইলগুলোর অবস্থা দেখায়।  
        যেমন: কোন ফাইল modified, added, deleted, untracked ইত্যাদি।
      </td>
    </tr>
    <tr>
      <td>3</td>
      <td><code>git clone &lt;URL&gt;</code></td>
      <td>Remote repository (যেমন GitHub) থেকে সম্পূর্ণ প্রজেক্ট local machine-এ নামিয়ে আনে।</td>
    </tr>
    <tr>
      <td>4</td>
      <td><code>git add</code></td>
      <td>
        Working directory থেকে ফাইলের পরিবর্তনগুলো staging area-তে পাঠায়, যাতে commit করা যায়।
      </td>
    </tr>
    <tr>
      <td>5</td>
      <td><code>git reset</code></td>
      <td>Staging area থেকে ফাইল সরিয়ে আবার working directory-তে পাঠায়।</td>
    </tr>
    <tr>
      <td>6</td>
      <td><code>git restore --staged file_name</code></td>
      <td>Staging area থেকে নির্দিষ্ট ফাইল remove করে, কিন্তু ফাইল delete করে না।</td>
    </tr>
    <tr>
      <td>7</td>
      <td><code>git restore file_name</code></td>
      <td>Local machine থেকে delete বা পরিবর্তিত ফাইল আগের অবস্থায় ফিরিয়ে আনে।</td>
    </tr>
    <tr>
      <td>8</td>
      <td><code>git commit -m "message"</code></td>
      <td>Staging area-তে থাকা পরিবর্তনগুলো permanently Git repository-তে সংরক্ষণ করে।</td>
    </tr>
    <tr>
      <td>9</td>
      <td><code>git reset HEAD~</code></td>
      <td>শেষ commit বাতিল করে ফাইলগুলো আবার working directory-তে নিয়ে আসে।</td>
    </tr>
    <tr>
      <td>10</td>
      <td><code>git reset --hard</code></td>
      <td>
        সব পরিবর্তন স্থায়ীভাবে মুছে ফেলে এবং আগের অবস্থায় ফিরিয়ে নেয়।
        (সতর্কতার সাথে ব্যবহার করতে হয়)
      </td>
    </tr>
    <tr>
      <td>11</td>
      <td><code>git rm file_name</code></td>
      <td>ফাইল delete করে এবং একই সাথে staging area-তে পাঠায়।</td>
    </tr>
    <tr>
      <td>12</td>
      <td><code>git rm -f file_name</code></td>
      <td>Modified থাকা ফাইল জোরপূর্বক delete করে এবং staging করে।</td>
    </tr>
    <tr>
      <td>13</td>
      <td><code>git rm --cached file_name</code></td>
      <td>ফাইল Git tracking থেকে সরায়, কিন্তু local machine-এ রেখে দেয়।</td>
    </tr>
    <tr>
      <td>14</td>
      <td><code>git rm -r folder_name</code></td>
      <td>পুরো একটি folder এবং তার ভেতরের সব ফাইল delete করে।</td>
    </tr>
    <tr>
      <td>15</td>
      <td><code>git branch</code></td>
      <td>Repository-তে থাকা সব branch-এর তালিকা দেখায়।</td>
    </tr>
    <tr>
      <td>16</td>
      <td><code>git branch branch_name</code></td>
      <td>নতুন একটি branch তৈরি করে।</td>
    </tr>
    <tr>
      <td>17</td>
      <td><code>git checkout branch_name</code></td>
      <td>এক branch থেকে অন্য branch-এ switch করে।</td>
    </tr>
    <tr>
      <td>18</td>
      <td><code>git merge branch_name</code></td>
      <td>অন্য একটি branch-এর পরিবর্তন বর্তমান branch-এ যুক্ত করে।</td>
    </tr>
    <tr>
      <td>19</td>
      <td><code>git push origin branch_name</code></td>
      <td>Local branch-এর commit গুলো Remote repository (GitHub)-এ পাঠায়।</td>
    </tr>
    <tr>
      <td>20</td>
      <td><code>git fetch</code></td>
      <td>
        Remote repository থেকে নতুন commit ও branch-এর তথ্য আনে,
        কিন্তু Local branch-এর সাথে merge করে না।
      </td>
    </tr>
    <tr>
      <td>21</td>
      <td><code>git pull</code></td>
      <td>
        Remote repository থেকে update এনে Local branch-এর সাথে merge করে।
        (git fetch + git merge)
      </td>
    </tr>
    <tr>
      <td>22</td>
      <td><code>git log</code></td>
      <td>commit history দেখাবে</td>
    </tr>
    <tr>
      <td>23</td>
      <td><code>git log --oneline</code></td>
      <td>প্রতিটি commit-এর সংক্ষিপ্ত hash এবং message দেখা যাবে</td>
    </tr>
    <tr>
      <td>24</td>
      <td><code>git checkout commit_hash </code></td>
      <td>নির্দিষ্ট commit-এর state-এ যেতে</td>
    </tr>
    <tr>
      <td>25</td>
      <td><code>git show commit_hash </code></td>
      <td>শুধু commit-এর পরিবর্তনগুলো দেখতে চাওয়া</td>
    </tr>
  </tbody>
</table>



| Status | Meaning        |
| ------ | -------------- |
| `A`    | Added to stage |
| `M`    | Modified       |
| `D`    | Deleted        |
| `R`    | Renamed        |
| `U`    | Unmerged       |
