# Bandit Level 4 → Level 5

## Task
[-> link](https://overthewire.org/wargames/bandit/bandit5.html)

The password for the next level is stored in the only human-readable file in the inhere directory.
Tip: if your terminal is messed up, try the “reset” command.

## Solution

```shell
ssh bandit4@bandit.labs.overthewire.org -p 2220  # (with password 'xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq')
cd inhere && for file in *; do if [ -f "${file}" ]; then cat -- "${file}" && printf "\n\n"; fi; done
```

## Result

```text
<Э�����4���b�y����ͻQ�Ov�N+Ď

����:�|�Y|fEHUv�#�����P��}

O�9�pJ
      �(�g�%�j~6��ɹ���l���9�

2R謡g���B�Ef�>c���ڂ~E9&��n

�J��3�c��ـ�{~����hI�x.�d�k>

�

dgy��Bp�7�
������6�s�� Z70�


��MW�� �jN<�a�L�Lj=1���

6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG


�T�|��6��Դ9�(��
               ^�����*��8

E�b�Ҍ9L��'R�U��R�5���閭
                       ��
```

We've got password `6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG`!
