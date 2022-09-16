# Proposal Process

The primary purpose of this repository is to provide visibility into the feature
development process for HLSL and solicit feedback from the wider community.
Despite the openness of this process there are three significant caveats that
should be noted:

1. Final decisions about what features are included or excluded from HLSL are
  made by the MSFT HLSL Team.
2. This process cannot be used for features that require Shader Model changes
  because Shader Model collaboration with hardware vendors occurs in private
  under NDA.
3. Some HLSL features may not go through this process, and may be kept secret
  during development. We will try to restrict this only to features that require
  NDAs with hardware vendors, but that may not always be the reason.

Feature proposals from outside the HLSL team will be interpreted as requests,
and may be considered or rejected based on team and release priorities. You
should not create a pull request against this repository if you're not committed
to at least making a best effort to navigate the process as described below.

If you want to request a feature but not get involved in the process, the best
way to request features for HLSL is to file GitHub issues rather than creating
pull requests against this repository.

This process draws heavily from
[Rust's RFC process](https://github.com/rust-lang/rfcs), and from
[Swift's Evolution process](https://github.com/apple/swift-evolution/), and is
further tweaked to align with the HLSL team's goals and priorities.

## Proposing a Feature

By far the best way for an external contributor to propose a feature is through
GitHub issues. If you can't be deterred from writing a proposal yourself you
must find a member of the HLSL team to act as a _Sponsor_ for the change. The
_Sponsor_ is responsible for tracking and helping change proposals through the
proposal life cycle.

All feature proposals are evaluated against the goals for the next HLSL language
revision. The goals for the upcoming HLSL language version can be found
[here](HLSL202x.md).

## Proposal Lifecycle

Draft proposals are first provided as pull requests. They should be written
following one of the templates in the `proposals/templates` directory.

Proposals that follow the most simplified path from idea to feature will move
through the following states in order:

* **Under Consideration** - All proposed features start in this state. While
  under consideration features are reviewed by members of the HLSL team and
  feedback is solicited from users and hardware vendors.

* **Under Review** - If a feature is deemed to be in alignment with the release
  goals, and of value to the community a feature may be promoted to being under
  review. During this time, a feature specification must be drafted, revised,
  and accepted.

* **Accepted** - Once a feature is accepted it becomes a planned feature for the
  release. At this time changes to enable the feature under the new language
  mode can begin landing in the HLSL compiler. The Accepted state does not mean
  the feature will ship in the planned release. There are a variety of reasons
  why features may not make the final release, but it does signify an intent to
  bring the feature into the release.

* **Completed** - Once a feature is fully implemented in the main compiler
  branch under the appropriate language version, the proposal completed.

Additionally feature proposals may end up in the **Rejected** or **Deferred**
states.

**Rejected** features are features that will not be included in HLSL. All
rejected features will be appended with a detailed reasoning explaining the
rationale behind why the feature was rejected.

**Deferred** features can occur for a variety of reasons. Features that are
deferred may be provided with some justification for the deferral although the
requirements for justification are not high and could be as simple as
"insufficient resources".
